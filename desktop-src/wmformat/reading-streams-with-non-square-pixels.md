---
title: Lesen Streams mit nicht quadratischen Pixeln
description: Lesen Streams mit nicht quadratischen Pixeln
ms.assetid: 32114c81-cb78-43de-9ea7-f210056f5aab
keywords:
- Windows Medienformat-SDK, Lesen von Videostreams
- Windows Medienformat-SDK, Videostreams
- Windows Medienformat-SDK, nicht quadratische Pixel
- Windows Medienformat-SDK, Pixel (nicht quadratisch)
- Advanced Systems Format (ASF), Lesen von Videostreams
- ASF (Advanced Systems Format), Lesen von Videostreams
- Advanced Systems Format (ASF), Videostreams
- ASF (Advanced Systems Format), Videostreams
- Advanced Systems Format (ASF), nicht quadratische Pixel
- ASF (Advanced Systems Format), nicht quadratische Pixel
- Advanced Systems Format (ASF), Pixel (nicht quadratisch)
- ASF (Advanced Systems Format), Pixel (nicht quadratisch)
- Lesen von Videostreams
- Videostreams,Lesen
- Videostreams, nicht quadratische Pixel
- Nicht-Quadratpixel
- Pixel (nicht quadratisch)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9173c7b5dca81f11a6e35afafe30efa33d86c604adcadb59a51b17ab8130422c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117846027"
---
# <a name="reading-streams-with-non-square-pixels"></a>Lesen Streams mit nicht quadratischen Pixeln

Leseranwendungen, die nicht quadratische Pixel ordnungsgemäß verarbeiten müssen, sollten sowohl die Attribute auf Streamebene im ASF-Header als auch die Dateneinheitserweiterungen in jedem Beispiel untersuchen. Es gibt zwei Fälle, in denen das Ausgaberechteck angepasst werden muss, um nicht quadratische Pixel zu kompensieren.

Wenn der Quellinhalt von einem Gerät wie einer DV-Kamera (digitales Video) mit nicht quadratischen Pixeln im CCD erfasst wurde, muss eine Readeranwendung ihr Videoausgaberechteck so anpassen, dass das Bild ordnungsgemäß auf einem Computermonitor mit Quadratpixeln angezeigt wird.

Wenn Ihre Readeranwendung Videos ausgibt, die auf einem NTSC-Fernsehgerät abgespielt werden, z. B. über eine S-Video-Out-Verbindung auf der Grafikkarte, müssen Sie das Videorechteck so anpassen, dass das Bild ordnungsgemäß auf den nicht quadratischen Pixeln des Fernsehgeräts angezeigt wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**So lesen und schreiben Sie Streams mit nicht quadratischen Pixeln**](to-read-and-write-video-streams-with-non-square-pixels.md)
</dt> </dl>

 

 




