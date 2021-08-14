---
description: X3DAudio ist eine API, die mit XAudio2 verwendet wird, um Sound im 3D-Raum zu positionieren, um die Töne zu erzeugen, die von einem Punkt im Raum relativ zur Position der Kamera kommen.
ms.assetid: 1638e848-4186-5dea-18e8-5369eee544ae
title: Übersicht über X3DAudio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2eb39239027bf8c7387fbe4cb25b80cef88bb241b74facf0b7bd7ee35c77965b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118962549"
---
# <a name="x3daudio-overview"></a>Übersicht über X3DAudio

X3DAudio ist eine API, die mit [XAudio2](programming-guide.md) verwendet wird, um Sound im 3D-Raum zu positionieren, um die Töne zu erzeugen, die von einem Punkt im Raum relativ zur Position der Kamera kommen. Insbesondere titel, die 3D-Szenen verwenden, möchten X3DAudio verwenden. Sounds, die keine 3D-Positionierung erfordern, z. B. 3D-Töne oder nicht positionierte Umgebungssounds, umgehen X3DAudio möglicherweise vollständig.

## <a name="listeners-and-emitters"></a>Listener und Emitter

Zum Verwalten von Sounds im 3D-Raum verwendet X3DAudio die Konzepte von *Listenern* und *Emittern.* Listener und Emitter stellen die Position des 3D-Sounds und den Punkt dar, von dem diese Töne stammen.

-   Ein Listener wird als Punkt im Raum und als Ausrichtung definiert. Es ist die Position, an der der Sound gehört *wird.* Die Position und Ausrichtung des Listeners ist im Allgemeinen mit der Position und Ausrichtung der Kamera identisch. Dies gilt unabhängig davon, ob ein Titel eine Perspektive der ersten oder dritten Person verwendet. Die Position des Listeners wird in Weltkoordinaten ausgedrückt. Es ist wichtig zu beachten, dass  die Position des Listeners relativ zu einem Emitter bestimmt, wie die endgültigen Sprechervolumen berechnet werden.
-   Ein Emitter wird als ein (oder mehrere) Punkte im Raum definiert, aus dem ein Sound *stammt.* Die Position des Emitters kann an einer beliebigen Stelle im 3D-Raum sein. Wie ein Listener wird die Position eines Emitters in Weltkoordinaten ausgedrückt. Die Position des Emitters relativ *zum* Listener bestimmt, wie die endgültigen Sprechervolumes berechnet werden.
-   X3DAudio verwendet linkshändige Koordinaten. Um mit rechtshändigen Koordinaten zu verwenden, müssen Entwickler das .z-Element der Elemente "OrientTop", "OrientFront", "Position" und "Velocity" von X3DAUDIO LISTENER und \_ X3DAUDIO \_ EMITTER negieren.

Zusätzlich zur Position können Listener und Emitter Geschwindigkeiten enthalten. Im Gegensatz zu einer 3D-Rendering-Engine verwendet X3DAudio nur die Geschwindigkeit, um Dopplereffekte zu berechnen (es wird nicht zum Berechnen der Position verwendet).

Weitere Informationen zu Listenern und Emittern finden Sie in den Referenzthemen [**zur X3DAUDIO \_ LISTENER-**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_listener) und [**X3DAUDIO \_ EMITTER-Struktur.**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_emitter)

## <a name="using-x3daudio-with-xaudio2"></a>Verwenden von X3DAudio mit XAudio2

Verwenden Sie für alle Interaktionen zwischen X3DAudio und XAudio2 die folgenden X3DAudio-Funktionen.

-   [**X3DAudioInitialize**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudioinitialize)

    Rufen Sie die [**X3DAudioInitialize-Funktion auf,**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudioinitialize) um X3DAudio zu initialisieren. In der Regel müssen Sie **X3DAudioInitialize** nur einmal während der Lebensdauer eines Spiels aufrufen, es sei denn, die Sprecherkonfiguration wird geändert.

-   [**X3DAudioCalculate**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudiocalculate)

    Nachdem Sie X3DAudio initialisiert haben, können Sie die Lautstärke und andere Werte für einen bestimmten Sound bestimmen, indem Sie den Emitter des Sounds und den Listener an die [**X3DAudioCalculate-Funktion**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudiocalculate) übergeben. Die von **X3DAudioCalculate** berechneten Werte können dann entsprechend den an die Funktion übergebenen Flags auf XAudio2-Stimmen oder -Effekte angewendet werden. Sie können von X3DAudio berechnete Volumen- und Tonhöhenwerte mit den Methoden [**IXAudio2Voice::SetOutputMatrix**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputmatrix) und [**IXAudio2SourceVoice::SetFrequencyRatio**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-setfrequencyratio) auf eine Stimme anwenden. Andere von X3DAudio berechnete Werte müssen [](/windows/desktop/api/xaudio2fx/nf-xaudio2fx-xaudio2createreverb) mithilfe der [**IXAudio2Voice::SetEffectParameters-Methode**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectparameters) auf einen Halleffekt angewendet werden.

Ein schrittweises Beispiel für die Verwendung von X3DAudio mit XAudio2 finden Sie unter [How to: Integrate X3DAudio with XAudio (Integrieren von X3DAudio in XAudio).](how-to--integrate-x3daudio-with-xaudio2.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[X3DAudio](x3daudio.md)
</dt> </dl>

 

 
