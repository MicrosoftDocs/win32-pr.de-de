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
# <a name="adding-an-information-chunk"></a>Hinzufügen eines Informations Blocks

Wenn Sie zusätzlich zu Audioinformationen und Videos Weitere Informationen in Ihre Anwendung einschließen müssen, können Sie Informationsblöcke erstellen und in eine Aufzeichnungsdatei einfügen. Informationsblöcke können mehrere Arten von Informationen enthalten, einschließlich der Details eines Copyright Hinweises, der Identifizierung der Videoquelle oder externer Zeit Steuerungsinformationen. Im folgenden Beispiel werden die Informationen zur externen Zeitangabe a SMPTE (Society of Motion Picture and TV Engineers) Zeitcode in einem Informationsblock gespeichert und mithilfe des [**capflesetinfochunk**](/windows/desktop/api/Vfw/nf-vfw-capfilesetinfochunk) -Makros in eine Aufzeichnungsdatei eingefügt.


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



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden der Video Erfassung](using-video-capture.md)
</dt> </dl>

 

 




