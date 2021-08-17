---
title: Hinzufügen eines Informationsblöckes
description: Hinzufügen eines Informationsblöckes
ms.assetid: ebba5079-1f67-4236-9260-e36ff72ad51c
keywords:
- capFileSetInfoChunk-Makro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 420181fd0da326ebf3ccc6f921e55161c2005d17c3f8713cd104481147b40f1b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119145133"
---
# <a name="adding-an-information-chunk"></a>Hinzufügen eines Informationsblöckes

Wenn Sie neben Audio und Video weitere Informationen in Ihre Anwendung aufnehmen müssen, können Sie Informationsblöcke erstellen und in eine Aufzeichnungsdatei einfügen. Informationsblöcke können verschiedene Arten von Informationen enthalten, einschließlich der Details eines Urheberrechtshinweises, der Identifizierung der Videoquelle oder externer Zeitsteuerungsinformationen. Im folgenden Beispiel werden externe Zeitsteuerungsinformationen in einem SMPTE-Zeitcode (Society of Motion Picture and Tv Engineers) in einem Informationsblöcke gespeichert und mithilfe des Makros [**capFileSetInfoChunk**](/windows/desktop/api/Vfw/nf-vfw-capfilesetinfochunk) einer Erfassungsdatei hinzugefügt.


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

[Verwenden von Video capture](using-video-capture.md)
</dt> </dl>

 

 




