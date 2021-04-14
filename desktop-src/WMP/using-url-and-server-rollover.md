---
title: Verwenden von URL-und Serverrollover
description: Verwenden von URL-und Serverrollover
ms.assetid: d0d15b1c-5631-486e-8490-b85ec51bd355
keywords:
- Windows Media Metadatei-Wiedergabelisten, URL-Rollover
- Wiedergabelisten, URL-Rollover
- Metadatei-Wiedergabelisten, URL-Rollover
- Windows Media Metadatei-Wiedergabelisten, Serverrollover
- Wiedergabelisten, Serverrollover
- Metadatei-Wiedergabelisten, Serverrollover
- Windows Media Metadatei-Wiedergabelisten, Protokollrollover
- Wiedergabelisten, Protokollrollover
- Metadatei-Wiedergabelisten, Protokollrollover
- Windows Media Player, URL-Rollover
- Windows Media Player, Serverrollover
- Windows Media Player, Protokollrollover
- URL-Rollover
- Serverrollover
- Protokollrollover
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: eae38e81f8ae23199628e543f65f2766491f1a2a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310168"
---
# <a name="using-url-and-server-rollover"></a><span data-ttu-id="94b4e-118">Verwenden von URL-und Serverrollover</span><span class="sxs-lookup"><span data-stu-id="94b4e-118">Using URL and Server Rollover</span></span>

<span data-ttu-id="94b4e-119">Mithilfe von Metadatei-Wiedergabelisten können Sie ein automatisches Rollback zu alternativen Inhalts Quellen bereitstellen, wenn auf einen Stream nicht zugegriffen oder wiedergegeben werden kann.</span><span class="sxs-lookup"><span data-stu-id="94b4e-119">You can use metafile playlists to provide a means of automatically rolling over to alternate content sources when a stream cannot be accessed or played.</span></span> <span data-ttu-id="94b4e-120">Mit dieser Rollover-Methode können Sie Quellen desselben Inhalts auf unterschiedlichen Servern oder unterschiedlichen Server Typen angeben.</span><span class="sxs-lookup"><span data-stu-id="94b4e-120">You can use this rollover method to specify sources of the same content on different servers or different types of servers.</span></span> <span data-ttu-id="94b4e-121">Sie können z. b. eine erste Alternative auf einem anderen Windows Media-Server angeben.</span><span class="sxs-lookup"><span data-stu-id="94b4e-121">You can, for example, specify a first alternate on a different Windows Media server.</span></span> <span data-ttu-id="94b4e-122">Wenn diese Inhalte nicht wiedergegeben werden können, kann der Client ein Rollback auf eine zweite Alternative auf einem Webserver ausführen.</span><span class="sxs-lookup"><span data-stu-id="94b4e-122">If that content fails to play, the client can roll over to a second alternate on a web server.</span></span> <span data-ttu-id="94b4e-123">Windows Media Player versucht automatisch, gemäß seinen Windows Media-Eigenschafts Einstellungen ein Rollback auf verschiedene Protokolle auszuführen, bevor die Rollover-URLs in der Wiedergabeliste ausprobiert werden.</span><span class="sxs-lookup"><span data-stu-id="94b4e-123">Windows Media Player automatically tries to roll over to different protocols according to its Windows Media property settings before trying the rollover URLs in the playlist.</span></span>

<span data-ttu-id="94b4e-124">Legen Sie Server-und Protokollrollover fest, indem Sie mehrere **ref** -Elemente nacheinander innerhalb eines **Eintrags** Elements platzieren.</span><span class="sxs-lookup"><span data-stu-id="94b4e-124">Set server and protocol rollover by placing multiple **REF** elements in succession within one **ENTRY** element.</span></span> <span data-ttu-id="94b4e-125">Jedes **ref** -Element gibt einen alternativen Speicherort oder ein alternatives Protokoll für eine Mediendatei oder einen Datenstrom an.</span><span class="sxs-lookup"><span data-stu-id="94b4e-125">Each **REF** element specifies an alternate location or protocol for a media file or stream.</span></span>

<span data-ttu-id="94b4e-126">Beispielcode</span><span class="sxs-lookup"><span data-stu-id="94b4e-126">Example Code</span></span>


```XML
<!--Server and protocol rollover is set for the file Rollover.wma.-->
<ASX version="3.0">
    <TITLE>MyServer Rollover</TITLE>
   <ENTRY>
      <REF HREF="mms://Server1.proseware.com/Path/Rollover.wma"/>
      <REF HREF="mms://Server2.proseware.com/Path/Rollover.wma"/>
      <REF HREF="mms://Server3.proseware.com/Path/Rollover.wma"/>
      <REF HREF="https://www.proseware.com/Path/Rollover.wma"/>
   </ENTRY>
</ASX>

```



## <a name="related-topics"></a><span data-ttu-id="94b4e-127">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="94b4e-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="94b4e-128">**Erstellen von Metafile-Wiedergabelisten**</span><span class="sxs-lookup"><span data-stu-id="94b4e-128">**Creating Metafile Playlists**</span></span>](creating-metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="94b4e-129">**Verwenden von Metafile-Wiedergabelisten**</span><span class="sxs-lookup"><span data-stu-id="94b4e-129">**Using Metafile Playlists**</span></span>](using-metafile-playlists.md)
</dt> </dl>

 

 




