---
title: Video (Windows Media Player SDK)
description: Video
ms.assetid: 3c654494-19b5-401e-bed8-02f7cc7d7f4e
keywords:
- Windows Media Player Mobile Skins,Video
- Skins,Video
- Referenz für Skins,Video
- Video in Skins, Informationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c116be7371191780d4939e15c99b30437c895adb31de6d207e120be9225af628
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117931387"
---
# <a name="video-windows-media-player-sdk"></a>Video (Windows Media Player SDK)

Mit einer Videoanzeige kann der Benutzer digitale Videodateien anzeigen. Der Videoanzeigebereich ist nur sichtbar, wenn das Video abspielt oder angehalten wird. Wenn Sie Ihre Skin entwerfen, sollten Sie Platz im Hintergrundbild reservieren, um die Videoanzeige zu enthalten. Wenn dies nicht der Fall ist, überlagert sich die Videoanzeige möglicherweise selbst über alle sichtbaren Artefakte, z. B. die Hintergrunddatei, Schaltflächen und Trackbars, die den Benutzer davon abhält, die Steuerelemente auf Ihrer Skin zu verwenden.

Der Abschnitt Video der Skindefinitionsdatei muss mit dieser Zeile beginnen:


```C++
[ Video ]

```



Anschließend müssen Sie eine Zeile hinzufügen, die die Position und Größe des Videoanzeigebereichs in Ihrer Skin angibt.


```C++
0,38,240,172

```



Sie können die folgende Vorlage für den Abschnitt Video Ihrer Skindefinitionsdatei verwenden:


```C++
//  <Location>
//  ----------

```



Die folgenden Abschnitte enthalten weitere Details.

-   [Videospeicherort](video-location.md)
-   [Videobildquelle](video-image-source.md)
-   [Videogröße](video-size.md)
-   [Abschnitt "Beispielvideo"](sample-video-section.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Skin-Referenz**](skin-reference.md)
</dt> </dl>

 

 




