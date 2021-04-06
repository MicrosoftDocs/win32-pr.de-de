---
title: Rich-Media-Streaming
description: Rich-Media-Streaming
ms.assetid: 3a48ee9a-5bf8-4cd0-9eed-07ec6da0f578
keywords:
- Windows Media Player, webbasierte Präsentationen
- Windows Media Player-Objektmodell, webbasierte Präsentationen
- Objektmodell, webbasierte Präsentationen
- Windows Media Player Mobile, webbasierte Präsentationen
- Windows Media Player ActiveX-Steuerelement, webbasierte Präsentationen
- Windows Media Player Mobile ActiveX-Steuerelement, webbasierte Präsentationen
- ActiveX-Steuerelement, webbasierte Präsentationen
- Windows Media Player, Rich-Media-Streaming
- Windows Media Player-Objektmodell, Rich-Media-Streaming
- Objektmodell, Rich-Media-Streaming
- Windows Media Player Mobile, Rich-Media-Streaming
- Windows Media Player ActiveX-Steuerelement, Rich-Media-Streaming
- Windows Media Player Mobile ActiveX-Steuerelement, Rich-Media-Streaming
- ActiveX-Steuerelement, Rich-Media-Streaming
- Webbasierte Präsentationen, Rich-Media-Streaming
- Erstellen von webbasierten Präsentationen, Rich-Media-Streaming
- Rich-Media-Streaming
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54b454ef62f5f5aaaf424598d55d85c03684538c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103712714"
---
# <a name="rich-media-streaming"></a><span data-ttu-id="0407e-120">Rich-Media-Streaming</span><span class="sxs-lookup"><span data-stu-id="0407e-120">Rich Media Streaming</span></span>

<span data-ttu-id="0407e-121">Komplexe Webseiten enthalten viele verschiedene Komponenten, die normalerweise separat übertragen werden.</span><span class="sxs-lookup"><span data-stu-id="0407e-121">Complex webpages contain many different components that are normally transferred separately.</span></span> <span data-ttu-id="0407e-122">Bei einer langsamen Verbindung werden solche Seiten jeweils nacheinander angezeigt, und es kann einige Minuten dauern, bis Sie vollständig angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="0407e-122">On a slow connection, such pages display one piece at a time and may take several minutes to display completely.</span></span> <span data-ttu-id="0407e-123">Dadurch wird möglicherweise verhindert, dass Webseiten mit digitalen Medien synchronisiert werden.</span><span class="sxs-lookup"><span data-stu-id="0407e-123">This may prevent you from effectively synchronizing webpages with your digital media.</span></span> <span data-ttu-id="0407e-124">Die Lösung für dieses Problem ist das umfangreiche Medien Streaming. Dies bedeutet, dass Sie Ihre Webseiten zu Ihrem Digital Media-Stream hinzufügen, sodass Sie zur gleichen Zeit wie die Audiodaten oder Videodaten bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="0407e-124">The solution to this problem is rich media streaming, which means adding your webpages to your digital media stream so that they are delivered at the same time as the audio or video data.</span></span>

<span data-ttu-id="0407e-125">Rich-Media-Streaming verwendet ein einfaches framesetlayout und verhält sich genau wie das normale URL-Flipping.</span><span class="sxs-lookup"><span data-stu-id="0407e-125">Rich media streaming uses a simple frameset layout and behaves exactly like normal URL flipping.</span></span> <span data-ttu-id="0407e-126">Ebenso wie beim URL-Flipping werden die in digitale Medienströme eingebetteten URL-Skript Befehle verwendet, um den Inhalt im Zielframe anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="0407e-126">Just as in URL flipping, URL script commands embedded in digital media streams are used to display the content in the target frame.</span></span> <span data-ttu-id="0407e-127">Anstatt auf Seiten im Web zu verweisen, werden die URL-Skript Befehle jedoch von der Windows Media Player 9-Serie oder höher verwendet, um auf Dateien im Internet Explorer-Cache zuzugreifen, in denen der übertragene HTML-Inhalt beim Empfang platziert wird.</span><span class="sxs-lookup"><span data-stu-id="0407e-127">Instead of pointing to pages on the Web, however, the URL script commands are used by Windows Media Player 9 Series or later to access files in the Internet Explorer cache where the streamed HTML content is placed as it is received.</span></span> <span data-ttu-id="0407e-128">Ebenso wie beim normalen URL-Flipping können Sie Ereignishandler schreiben, die auf diese URL-Skript Befehle reagieren, oder Sie können das Windows Media Player-Steuerelement automatisch verarbeiten lassen.</span><span class="sxs-lookup"><span data-stu-id="0407e-128">Just as with normal URL flipping, you can write event handlers that respond to these URL script commands, or you can let the Windows Media Player control handle everything automatically.</span></span>

> [!Note]  
> <span data-ttu-id="0407e-129">Alle HTML-Inhalte, die über das Rich-Media-Streaming bereitgestellt werden, werden in der Internet Sicherheitszone wiedergegeben und unterliegen den Browser Sicherheitseinstellungen des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="0407e-129">Any HTML content delivered through rich media streaming is played back in the Internet security zone, and is subject to the user's browser security settings.</span></span>

 

<span data-ttu-id="0407e-130">Weitere Informationen zum Erstellen von Rich-Media-Präsentationen finden Sie im Windows Media-Format 9 oder höher und im Windows Media Encoder 9-Serien-SDK.</span><span class="sxs-lookup"><span data-stu-id="0407e-130">For more information on creating rich media presentations, see the Windows Media Format 9 Series or later SDK and the Windows Media Encoder 9 Series SDK.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0407e-131">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="0407e-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0407e-132">**Erstellen von Web-Based Präsentationen**</span><span class="sxs-lookup"><span data-stu-id="0407e-132">**Creating Web-Based Presentations**</span></span>](creating-web-based-presentations.md)
</dt> <dt>

[<span data-ttu-id="0407e-133">**Verwenden von Skripts zum Steuern von URL-Flipping**</span><span class="sxs-lookup"><span data-stu-id="0407e-133">**Using Script to Control URL Flipping**</span></span>](using-script-to-control-url-flipping.md)
</dt> </dl>

 

 




