---
title: Anpassen von Geschwindigkeit, Volume und Zoom
description: Anpassen von Geschwindigkeit, Volume und Zoom
ms.assetid: 16cfbf86-911e-4cf3-9640-69fffc09c1ed
keywords:
- Mciwndsetspeed-Makro
- Mciwndgetspeed-Makro
- Mciwndsetvolume-Makro
- Mciwndgetvolume-Makro
- Mciwndsetzoom-Makro
- Mciwndgetzoom-Makro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f02b1e14a5153e279e3cfdf6989beade31cf6f3e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388350"
---
# <a name="adjusting-speed-volume-and-zoom"></a>Anpassen von Geschwindigkeit, Volume und Zoom

Die Makros "Geschwindigkeit", "Volume" und "Zoom" stellen die Funktionalität der Befehle " **View**", " **Volume**" und " **Speed** " im mciwnd-Menü bereit. Die in diesem Abschnitt beschriebenen Makros werden im Allgemeinen mit Videos und anderen Geräten verwendet, die während der Wiedergabe Bilder anzeigen.

Einige Geräte unterstützen mehrere Wiedergabe Geschwindigkeitsänderungen. Sie können die Wiedergabegeschwindigkeit für diese Geräte mit dem [**mciwndsetspeed**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetspeed) -Makro festlegen. Dieses Makro definiert die Wiedergabegeschwindigkeit als 1000. Höhere Werte weisen auf schnellere Geschwindigkeiten hin. Niedrigere Werte weisen auf eine langsamere Geschwindigkeit hin.

Sie können die aktuelle Wiedergabegeschwindigkeit abrufen, indem Sie das [**mciwndgetspeed**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetspeed) -Makro verwenden. Dieses Makro verwendet dieselben Werte und denselben Bereich wie die von **mciwndsetspeed** verwendeten Werte.

Einige Geräte unterstützen volumeänderungen. Sie können das Volume anpassen oder festlegen, indem Sie das [**mciwndsetvolume**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetvolume) -Makro verwenden. Dieses Makro definiert die normale Volumeebene als 1000. Höhere Werte weisen auf lauter Volumes hin. Niedrigere Werte weisen auf ruhigere Volumes hin.

Sie können die aktuelle Volumeebene abrufen, indem Sie das [**mciwndgetvolume**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetvolume) -Makro verwenden. Dieses Makro verwendet dieselben numerischen Werte und denselben Bereich wie die von **mciwndsetvolume** verwendeten Werte.

Bei Geräten, die ein Wiedergabe Fenster verwenden, unterstützt mciwnd eine Zoomfunktion, mit der die Größe des Wiedergabe Bilds festgelegt wird. Sie können die Wiedergabe Bildgröße mit dem [**mciwndsetzoom**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetzoom) -Makro festlegen. Das Makro definiert die Wiedergabe Bildgröße neu, während gleichzeitig ein konstantes Seitenverhältnis für das Bild beibehalten wird. Der Zoomwert wird als Prozentsatz der ursprünglichen Bildgröße definiert. Daher stellt 100 die ursprüngliche Bildgröße dar, 50 gibt an, dass das angezeigte Bild eine halbe Originalgröße hat, und 200, dass das angezeigte Bild doppelt so groß wie die ursprüngliche Größe ist.

Sie können den aktuellen Zoomwert abrufen, indem Sie das [**mciwndgetzoom**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetzoom) -Makro verwenden. Dieses Makro verwendet dieselben Werte und denselben Bereich wie die von **mciwndsetzoom** verwendeten Werte.

> [!Note]  
> Die standardmäßigen MCI-CD-Audiodaten und Waveform-Audiotreiber unterstützen keine Volumen-oder Geschwindigkeitsänderungen.

 

 

 




