---
title: Video (Windows Media Player SDK)
description: Video
ms.assetid: 3c654494-19b5-401e-bed8-02f7cc7d7f4e
keywords:
- Windows Media Player Mobile Skins, Video
- Skins, Video
- Referenz für Skins, Video
- Video in Skins, Informationen zu
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb3d505acec3f6917c7ed3d182c656ff5e9f29f0
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "106340553"
---
# <a name="video-windows-media-player-sdk"></a>Video (Windows Media Player SDK)

Eine Videoanzeige ermöglicht dem Benutzer die Anzeige digitaler Videodateien. Der Anzeigebereich des Videos ist nur sichtbar, wenn das Video abgespielt oder angehalten wird. Wenn Sie Ihre Skin entwerfen, sollten Sie Platz im Hintergrundbild reservieren, um die Videoanzeige zu enthalten. Wenn Sie dies nicht tun, kann sich die Videoanzeige selbst über alle sichtbaren Grafiken, wie z. b. die Hintergrund Datei, Schaltflächen und trackbars, übernehmen, sodass der Benutzer die Steuerelemente auf der Skin nicht mehr bedienen kann.

Der Video Abschnitt der Skin-Definitionsdatei muss mit der folgenden Zeile beginnen:


```C++
[ Video ]

```



Anschließend müssen Sie eine Zeile hinzufügen, die den Speicherort und die Größe des Videoanzeige Bereichs in der Skin angibt.


```C++
0,38,240,172

```



Sie können die folgende Vorlage für den Video Abschnitt Ihrer Skin-Definitionsdatei verwenden:


```C++
//  <Location>
//  ----------

```



In den folgenden Abschnitten finden Sie weitere Informationen.

-   [Video Speicherort](video-location.md)
-   [Video Bildquelle](video-image-source.md)
-   [Video Größe](video-size.md)
-   [Beispiel für einen Video Abschnitt](sample-video-section.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Skin-Referenz**](skin-reference.md)
</dt> </dl>

 

 




