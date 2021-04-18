---
title: Lesen von Streams mit nicht quadratischen Pixeln
description: Lesen von Streams mit nicht quadratischen Pixeln
ms.assetid: 32114c81-cb78-43de-9ea7-f210056f5aab
keywords:
- Windows Media-Format-SDK, Lesen von Videostreams
- Windows Media-Format-SDK, Videostreams
- Windows Media-Format-SDK, nicht eckige Pixel
- Windows Media-Format-SDK, Pixel (ohne Quadrat)
- Advanced Systems Format (ASF), Lesen von Videostreams
- ASF (Advanced Systems Format), Lesen von Videostreams
- Advanced Systems Format (ASF), Videostreams
- ASF (Advanced Systems Format), Videostreams
- Advanced Systems Format (ASF), nicht quadratische Pixel
- ASF (Advanced Systems Format), nicht eckige Pixel
- Advanced Systems Format (ASF), Pixel (ohne Quadrat)
- ASF (Advanced Systems Format), Pixel (ohne Quadrat)
- Lesen von Videostreams
- Videostreams, lesen
- Videostreams, nicht quadratische Pixel
- nicht quadratische Pixel
- Pixel (nicht quadratisch)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecfc14019e9822aefedb7600adc4209317293b2f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106338223"
---
# <a name="reading-streams-with-non-square-pixels"></a>Lesen von Streams mit nicht quadratischen Pixeln

Reader-Anwendungen, die nicht quadratische Pixel ordnungsgemäß verarbeiten müssen, sollten sowohl die Attribute auf Streamebene im ASF-Header als auch die Dateneinheiten Erweiterungen in jedem Beispiel untersuchen. Es gibt zwei Fälle, in denen das Ausgabe Rechteck so angepasst werden muss, dass es nicht quadratische Pixel kompensiert.

Wenn der Quell Inhalt von einem Gerät, wie z. b. einer DV-Kamera (Digital Video), mit nicht quadratischen Pixeln in seinem CCD aufgezeichnet wurde, muss eine Reader-Anwendung das Videoausgabe Rechteck anpassen, damit das Bild auf einem Computermonitor mit quadratischen Pixeln ordnungsgemäß angezeigt wird.

Wenn die Reader-Anwendung Videos ausgibt, die auf einem NTSC-Fernsehgerät wiedergegeben werden, z. b. über eine e-Video-out-Verbindung auf der Grafikkarte, müssen Sie das Video Rechteck anpassen, damit das Bild auf den nicht quadratischen Pixeln des Fernseh ERS ordnungsgemäß angezeigt wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**So lesen und schreiben Sie Videostreams mit nicht quadratischen Pixeln**](to-read-and-write-video-streams-with-non-square-pixels.md)
</dt> </dl>

 

 




