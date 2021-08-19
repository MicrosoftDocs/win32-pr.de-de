---
description: X3DAudio ist eine API, die mit XAudio2 verwendet wird, um Sound im 3D-Raum zu positionieren, um die Vorstellung von Sound zu erzeugen, der von einem Punkt im Raum relativ zur Position der Kamera stammt.
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

X3DAudio ist eine API, die mit [XAudio2](programming-guide.md) verwendet wird, um Sound im 3D-Raum zu positionieren, um die Vorstellung von Sound zu erzeugen, der von einem Punkt im Raum relativ zur Position der Kamera stammt. Insbesondere Titel, die 3D-Szenen enthalten, möchten X3DAudio verwenden. Sounds, die keine 3D-Positionierung erfordern, z. B. Töne oder nicht positionierte Umgebungssounds, können X3DAudio vollständig umgehen.

## <a name="listeners-and-emitters"></a>Listener und Emitter

Um Sounds im 3D-Raum zu verwalten, verwendet X3DAudio die Konzepte von *Listenern* und *Emittern.* Listener und Emitter stellen die Position des hörenden 3D-Sounds und den Punkt dar, von dem diese Sounds stammen.

-   Ein Listener wird als Punkt im Raum und als Ausrichtung definiert. Dies ist die Position, an der der Sound *gehört* wird. Die Position und Ausrichtung des Listeners entspricht im Allgemeinen der Position und Ausrichtung der Kamera. Dies gilt unabhängig davon, ob ein Titel eine Perspektive einer Ersten Person oder einer Perspektive einer dritten Person verwendet. Die Position des Listeners wird in Weltkoordinaten ausgedrückt. Es ist wichtig zu beachten, dass es die Position des Listeners *relativ* zu einem Emitter ist, der bestimmt, wie die endgültigen Sprechervolumen berechnet werden.
-   Ein Emitter wird als ein (oder mehrere) Punkte im Raum definiert, von dem ein Sound *stammt.* Die Position des Emitters kann sich an einer beliebigen Stelle im 3D-Raum befinden. Wie ein Listener wird die Position eines Emitters in Weltkoordinaten ausgedrückt. Die Position des Emitters *relativ* zum Listener bestimmt, wie die endgültigen Lautsprechervolumen berechnet werden.
-   X3DAudio verwendet linkshändige Koordinaten. Um mit rechtshändigen Koordinaten zu verwenden, müssen Entwickler das .z-Element der Elemente "OrientTop", "OrientFront", "Position" und "Velocity" von X3DAUDIO \_ LISTENER und X3DAUDIO \_ EMITTER negieren.

Zusätzlich zur Position können Listener und Emitter die Geschwindigkeit einschließen. Im Gegensatz zu einer 3D-Rendering-Engine verwendet X3DAudio nur die Geschwindigkeit, um Dopplereffekte zu berechnen (sie wird nicht zum Berechnen der Position verwendet).

Weitere Informationen zu Listenern und Emittern finden Sie in den Referenzthemen [**zur X3DAUDIO \_ LISTENER-**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_listener) und [**X3DAUDIO \_ EMITTER-Struktur.**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_emitter)

## <a name="using-x3daudio-with-xaudio2"></a>Verwenden von X3DAudio mit XAudio2

Verwenden Sie für alle Interaktionen zwischen X3DAudio und XAudio2 die folgenden X3DAudio-Funktionen.

-   [**X3DAudioInitialize**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudioinitialize)

    Rufen Sie die [**X3DAudioInitialize-Funktion**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudioinitialize) auf, um X3DAudio zu initialisieren. In der Regel müssen Sie **X3DAudioInitialize** nur einmal während der Lebensdauer eines Spiels aufrufen, es sei denn, die Konfiguration des Sprechers wird geändert.

-   [**X3DAudioCalculate**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudiocalculate)

    Nachdem Sie X3DAudio initialisiert haben, können Sie die Lautstärke und andere Werte für einen bestimmten Sound bestimmen, indem Sie den Emitter des Sounds und den Listener an die [**X3DAudioCalculate-Funktion**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudiocalculate) übergeben. Die von **X3DAudioCalculate berechneten** Werte können dann entsprechend den an die Funktion übergebenen Flags auf XAudio2-Stimmen oder -Effekte angewendet werden. Mit den Methoden [**IXAudio2Voice::SetOutputMatrix**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputmatrix) und [**IXAudio2SourceVoice::SetFrequencyRatio**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-setfrequencyratio) können Sie von X3DAudio berechnete Volumen- und Tonhöhenwerte auf eine Stimme anwenden. Andere von X3DAudio berechnete Werte müssen mithilfe der [**IXAudio2Voice::SetEffectParameters-Methode**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectparameters) auf einen [**Halleffekt**](/windows/desktop/api/xaudio2fx/nf-xaudio2fx-xaudio2createreverb) angewendet werden.

Ein Schritt-für-Schritt-Beispiel für die Verwendung von X3DAudio mit XAudio2 finden Sie unter [Vorgehensweise: Integrieren von X3DAudio in XAudio.](how-to--integrate-x3daudio-with-xaudio2.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[X3DAudio](x3daudio.md)
</dt> </dl>

 

 
