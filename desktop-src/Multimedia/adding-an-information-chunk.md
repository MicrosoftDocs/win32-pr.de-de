---
title: Hinzufügen eines Informations Blocks
description: Hinzufügen eines Informations Blocks
ms.assetid: ebba5079-1f67-4236-9260-e36ff72ad51c
keywords:
- capflesetinfochunk-Makro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bacb99fb29e4b1882b4f257c428315f42ee3a360
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104206903"
---
# <a name="adding-an-information-chunk"></a><span data-ttu-id="046a5-104">Hinzufügen eines Informations Blocks</span><span class="sxs-lookup"><span data-stu-id="046a5-104">Adding an Information Chunk</span></span>

<span data-ttu-id="046a5-105">Wenn Sie zusätzlich zu Audioinformationen und Videos Weitere Informationen in Ihre Anwendung einschließen müssen, können Sie Informationsblöcke erstellen und in eine Aufzeichnungsdatei einfügen.</span><span class="sxs-lookup"><span data-stu-id="046a5-105">If you need to include other information in your application in addition to audio and video, you can create information chunks and insert them into a capture file.</span></span> <span data-ttu-id="046a5-106">Informationsblöcke können mehrere Arten von Informationen enthalten, einschließlich der Details eines Copyright Hinweises, der Identifizierung der Videoquelle oder externer Zeit Steuerungsinformationen.</span><span class="sxs-lookup"><span data-stu-id="046a5-106">Information chunks can contain several types of information, including the details of a copyright notice, identification of the video source, or external timing information.</span></span> <span data-ttu-id="046a5-107">Im folgenden Beispiel werden die Informationen zur externen Zeitangabe a SMPTE (Society of Motion Picture and TV Engineers) Zeitcode in einem Informationsblock gespeichert und mithilfe des [**capflesetinfochunk**](/windows/desktop/api/Vfw/nf-vfw-capfilesetinfochunk) -Makros in eine Aufzeichnungsdatei eingefügt.</span><span class="sxs-lookup"><span data-stu-id="046a5-107">The following example stores external timing information a SMPTE (Society of Motion Picture and Television Engineers) timecode in an information chunk and adds the chunk to a capture file using the [**capFileSetInfoChunk**](/windows/desktop/api/Vfw/nf-vfw-capfilesetinfochunk) macro.</span></span>


```C++
//  This example assumes the application controls 
//  the video source for preroll and postroll. 
CAPINFOCHUNK cic;
// . 
// . 
// . 
cic.fccInfoID = infotypeSMPTE_TIME;
cic.lpData = "00:20:30:12"; 
cic.cbData = strlen (cic.lpData) + 1;
capFileSetInfoChunk (hwndC, &cic); 
 
```



## <a name="related-topics"></a><span data-ttu-id="046a5-108">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="046a5-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="046a5-109">Verwenden der Video Erfassung</span><span class="sxs-lookup"><span data-stu-id="046a5-109">Using Video Capture</span></span>](using-video-capture.md)
</dt> </dl>

 

 




