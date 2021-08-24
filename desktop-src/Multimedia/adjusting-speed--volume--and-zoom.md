---
title: Anpassen von Geschwindigkeit, Lautstärke und Zoom
description: Anpassen von Geschwindigkeit, Lautstärke und Zoom
ms.assetid: 16cfbf86-911e-4cf3-9640-69fffc09c1ed
keywords:
- MCIWndSetSpeed-Makro
- MCIWndGetSpeed-Makro
- MCIWndSetVolume-Makro
- MCIWndGetVolume-Makro
- MCIWndSetZoom-Makro
- MCIWndGetZoom-Makro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbed63549683a92d457b9b91ac967ff9098235bf8d9cbd60b1ea332624886d9a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119808570"
---
# <a name="adjusting-speed-volume-and-zoom"></a>Anpassen von Geschwindigkeit, Lautstärke und Zoom

Die Makros für Geschwindigkeit, Lautstärke und Zoom stellen die Funktionen der Befehle **Ansicht,** **Volume** und **Geschwindigkeit** im Menü MCIWnd zur Verfügung. Die in diesem Abschnitt beschriebenen Makros werden im Allgemeinen mit Videos und anderen Geräten verwendet, die Bilder während der Wiedergabe anzeigen.

Einige Geräte unterstützen mehrere Änderungen der Wiedergabegeschwindigkeit. Sie können die Wiedergabegeschwindigkeit für diese Geräte mithilfe des [**Makros MCIWndSetSpeed**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetspeed) festlegen. Dieses Makro definiert die Wiedergabegeschwindigkeit als 1000. Höhere Werte weisen auf schnellere Geschwindigkeiten hin. Niedrigere Werte weisen auf langsamere Geschwindigkeiten hin.

Sie können die aktuelle Wiedergabegeschwindigkeit mithilfe des [**MCIWndGetSpeed-Makros**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetspeed) abrufen. Dieses Makro verwendet die gleichen Werte und den gleichen Bereich wie die von **MCIWndSetSpeed** verwendeten Werte.

Einige Geräte unterstützen Volumeänderungen. Sie können das Volume mithilfe des [**Makros MCIWndSetVolume**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetvolume) anpassen oder festlegen. Dieses Makro definiert die normale Volumeebene als 1000. Höhere Werte geben lautere Volumes an. Niedrigere Werte geben stillere Volumes an.

Sie können die aktuelle Volumeebene mithilfe des [**Makros MCIWndGetVolume**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetvolume) abrufen. Dieses Makro verwendet die gleichen numerischen Werte und den gleichen Bereich wie die von **MCIWndSetVolume.**

Für Geräte, die ein Wiedergabefenster verwenden, unterstützt MCIWnd eine Zoomfunktion, mit der die Größe des Wiedergabebilds bestimmt wird. Sie können die Größe des Wiedergabebilds mithilfe des [**Makros MCIWndSetZoom**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetzoom) festlegen. Das Makro definiert die Größe des Wiedergabebilds neu, während gleichzeitig ein konstantes Seitenverhältnis für das Bild beibehalten wird. Der Zoomwert wird als Prozentsatz der ursprünglichen Bildgröße definiert. Daher stellt 100 die ursprüngliche Bildgröße dar, 50 gibt an, dass das angezeigte Bild halb so groß wie die ursprüngliche Größe ist, und 200 gibt an, dass das dargestellte Bild doppelt so groß ist wie das originale Bild.

Sie können den aktuellen Zoomwert mithilfe des [**MCIWndGetZoom-Makros**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetzoom) abrufen. Dieses Makro verwendet die gleichen Werte und den gleichen Bereich wie die von **MCIWndSetZoom** verwendeten Werte.

> [!Note]  
> Die standardmäßigen MCI-CD-Audio- und Waveform-Audiotreiber unterstützen keine Volume- oder Geschwindigkeitsänderungen.

 

 

 




