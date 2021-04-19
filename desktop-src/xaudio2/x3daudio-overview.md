---
description: X3DAudio ist eine API, die mit XAudio2 verwendet wird, um Sound in 3D-Raum zu positionieren, um die Illusion von Sound zu erzeugen, der von einem Punkt im Raum relativ zur Position der Kamera stammt.
ms.assetid: 1638e848-4186-5dea-18e8-5369eee544ae
title: X3DAudio Übersicht
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff509b16556ee1932d2a2543ad5008ddcbaa5b92
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106366224"
---
# <a name="x3daudio-overview"></a>X3DAudio Übersicht

X3DAudio ist eine API, die mit [XAudio2](programming-guide.md) verwendet wird, um Sound in 3D-Raum zu positionieren, um die Illusion von Sound zu erzeugen, der von einem Punkt im Raum relativ zur Position der Kamera stammt. Insbesondere sollten Titel mit 3D-Szenen X3DAudio verwenden. Sounds, die keine 3D-Positionierung benötigen, wie z. b. Soundtracks oder nicht positionierte Ambient-Sounds, können X3DAudio vollständig umgehen.

## <a name="listeners-and-emitters"></a>Listener und Emitter

Zum Verwalten von Sounds im 3D-Raum nutzt X3DAudio die Konzepte der *Listener und* *Emitter*. Listener und Emitter stellen die Position eines beliebigen Hörens 3D-Sounds und den Punkt dar, von dem aus diese Sounds stammen.

-   Ein Listener ist als Punkt im Raum und als Ausrichtung definiert. Es ist die Position, an der der Sound *gehört*. Die Position und Ausrichtung des Listener sind im allgemeinen identisch mit der Position und Ausrichtung der Kamera. Dies gilt unabhängig davon, ob ein Titel eine Perspektive der ersten oder dritten Person verwendet. Die Position des Listers wird in globalen Koordinaten ausgedrückt. Es ist wichtig zu beachten, dass es sich um die Position des Listers in *Relation* zu einem Emitter handelt, der bestimmt, wie die endgültigen Lautsprecher Volumes berechnet werden.
-   Ein Emitter ist als ein oder mehrere Punkte im Raum definiert, aus denen ein Sound *stammt*. Die Position des Emitters kann sich an einer beliebigen Stelle im 3D-Bereich befinden. Wie ein Listener wird die Position eines emitters in Weltkoordinaten ausgedrückt. Es handelt sich um die Position des Emitters *relativ* zum Listener, der bestimmt, wie die abschließenden Lautsprecher Volumes berechnet werden.
-   X3DAudio verwendet linkshändige Koordinaten. Um mit rechts gerichteten Koordinaten zu verwenden, müssen Entwickler das. z-Element der Elemente orienttop, orientfront, Position und Velocity von X3DAUDIO \_ Listener und X3DAUDIO Emitter negieren \_ .

Neben der Position können Listener und Emitter auch Velocity enthalten. Anders als bei einem 3D-Renderingmodul verwendet X3DAudio nur Velocity zum Berechnen von Doppler Effekten (es wird nicht zum Berechnen der Position verwendet).

Weitere Informationen zu Listenern und Emittern finden Sie in den Referenz Themen [**X3DAUDIO \_ Listener**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_listener) und [**X3DAUDIO \_ Emitter**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_emitter) Structure.

## <a name="using-x3daudio-with-xaudio2"></a>Verwenden von X3DAudio mit XAudio2

Verwenden Sie für die gesamte Interaktion zwischen X3DAudio und XAudio2 die folgenden X3DAudio-Funktionen.

-   [**X3DAudioInitialize**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudioinitialize)

    Ruft die [**X3DAudioInitialize**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudioinitialize) -Funktion auf, um X3DAudio zu initialisieren. In der Regel müssen Sie **X3DAudioInitialize** nur einmal während der Lebensdauer eines Spiels aufzurufen, es sei denn, die Lautsprecher Konfiguration wird geändert.

-   [**X3DAudioCalculate**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudiocalculate)

    Nachdem Sie X3DAudio initialisiert haben, können Sie das Volume und andere Werte für einen bestimmten Sound ermitteln, indem Sie den Emitter des Sounds und den Listener an die [**X3DAudioCalculate**](/windows/desktop/api/x3daudio/nf-x3daudio-x3daudiocalculate) -Funktion übergeben. Die von **X3DAudioCalculate** berechneten Werte können dann nach Bedarf auf XAudio2 Stimmen oder Effekte angewendet werden, wenn Sie für die an die Funktion übergebenen Flags geeignet sind. Sie können von X3DAudio berechnete Volumen-und Tonwerte auf eine Stimme mit den Methoden [**IXAudio2Voice:: setoutputmatrix**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputmatrix) und [**IXAudio2SourceVoice:: setfrequencyratio**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-setfrequencyratio) anwenden. Andere durch X3DAudio berechnete Werte müssen mithilfe der [**IXAudio2Voice:: absffectparameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectparameters) -Methode auf einen [**Hall Effekt**](/windows/desktop/api/xaudio2fx/nf-xaudio2fx-xaudio2createreverb) angewendet werden.

Ein schrittweises Beispiel für die Verwendung von X3DAudio mit XAudio2 finden Sie unter Gewusst [wie: Integrieren von X3DAudio in xaudiodaten](how-to--integrate-x3daudio-with-xaudio2.md) .

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[X3DAudio](x3daudio.md)
</dt> </dl>

 

 
