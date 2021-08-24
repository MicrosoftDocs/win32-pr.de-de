---
description: Videocodierung mit temporaler Komprimierung
ms.assetid: df363017-97c5-45b0-b8a5-44ac73b7a0e7
title: Videocodierung mit temporaler Komprimierung (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10d663b0101353d9ce72dab45f0b85e594afcacf4aa8b8a99a6d61d2db0ae07d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119721350"
---
# <a name="video-encoding-with-temporal-compression-microsoft-media-foundation"></a>Videocodierung mit temporaler Komprimierung (Microsoft Media Foundation)

Um die höchstmöglichen Komprimierungsverhältnisse zu erzielen, verwenden die Windows Media Video-Codecs *die temporale Komprimierung.* Temporale Komprimierung ist ein Verfahren zum Reduzieren der komprimierten Videogröße, indem nicht jeder Frame als vollständiges Bild codiert wird. Die Frames, die vollständig codiert sind (z. B. ein statisches Bild), werden als *Keyframes bezeichnet.* Alle anderen Frames im Video werden durch Daten dargestellt, die die Änderung seit dem letzten Frame angeben. Diese Frames werden als *Deltaframes bezeichnet.*

Der Umfang der Komprimierung, der mithilfe der temporalen Komprimierung erreicht werden kann, hängt vom Inhalt ab. Wenn das Video statisch ist, ohne viel Bewegung oder andere Änderungen am Bild, können viele Deltaframes für jeden Keyframe erstellt werden. Je mehr Deltaframes verwendet werden, desto kleiner ist der codierte Videostream. Wenn das Video jedoch dynamisch ist, mit vielen Bewegungen oder sich ändernden Farben, ist der Vorteil der Verwendung der temporalen Komprimierung geringer.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Arbeiten mit Videos](workingwithvideo.md)
</dt> </dl>

 

 



