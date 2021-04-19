---
description: Video Codierung mit Temporaler Komprimierung
ms.assetid: df363017-97c5-45b0-b8a5-44ac73b7a0e7
title: Video Codierung mit Temporaler Komprimierung (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ee107d8bf6b1ef6b1700abff105b0bdb79f72f5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106360181"
---
# <a name="video-encoding-with-temporal-compression-microsoft-media-foundation"></a>Video Codierung mit Temporaler Komprimierung (Microsoft Media Foundation)

Um möglichst hohe Komprimierungs Verhältnisse zu erzielen, verwenden die Windows Media Video Codecs die *zeitliche Komprimierung*. Mit der temporalen Komprimierung wird die komprimierte Videogröße reduziert, indem die einzelnen Frames nicht als Ganzes Bild codiert werden Die Frames, die vollständig codiert werden (wie ein statisches Bild), werden als *Keyframes* bezeichnet. Alle anderen Frames im Video werden durch Daten dargestellt, die die Änderung seit dem letzten Frame angeben. Diese Frames werden als *Delta Frames* bezeichnet.

Der Umfang der Komprimierung, die mithilfe der temporalen Komprimierung erreicht werden kann, hängt vom Inhalt ab. Wenn das Video ohne großen Bewegungs Aufwand oder anderen Änderungen im Bild statisch ist, können für jeden Keyframe viele Delta Rahmen erstellt werden. Welche weiteren Delta Rahmen verwendet werden, desto kleiner ist der codierte Videostream. Wenn das Video jedoch dynamisch ist, aber viel Bewegung oder Farben hat, ist der Vorteil der Verwendung der temporalen Komprimierung geringer.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Arbeiten mit Videos](workingwithvideo.md)
</dt> </dl>

 

 



